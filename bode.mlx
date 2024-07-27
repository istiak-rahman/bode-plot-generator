% Define the transfer function coefficients
numerator_coefficients = [434.78, 1317.2622, 131738340];  % 434.78*(s^2 + 3.03s + 3.03e05)
denominator_coefficients = [1, 7.378, 7.378e05, 0, 0];  % s^2*(s^2 + 7.378s + 7.378e05)
 
% Define the transfer function
sys = tf(numerator_coefficients, denominator_coefficients);

% Define the frequency range
freq_range = linspace(100, 1000, 1000);  % 100 to 1000 rad/sec

% Get the frequency response of the system
[mag, phase, w] = bode(sys, freq_range);

% Plot the magnitude Bode plot
figure;
subplot(2, 1, 1);
semilogx(w, 20*log10(squeeze(mag)));  % Use squeeze to remove singleton dimensions
ylabel('Magnitude (dB)');
grid on;

% Plot the phase Bode plot
subplot(2, 1, 2);
semilogx(w, squeeze(phase));  % Use squeeze to remove singleton dimensions
xlabel('Frequency (rad/sec)');
ylabel('Phase (degrees)');
grid on;

% Set y-axis ticks for the phase plot
yticks(subplot(2, 1, 2), -180:45:0);
ylim(subplot(2, 1, 2), [-180, 0]);

% Adjust figure properties
sgtitle('Applied Torque to Motor Shaft Position');



