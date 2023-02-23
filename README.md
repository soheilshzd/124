# 124

theta = linspace(0,2*pi,100);
radius = 2; % set the radius of the circle
x = radius*cos(theta);
y = radius*sin(theta);
plot(x,y)



x1 = 1; % x-coordinate of starting point
y1 = 2; % y-coordinate of starting point
x2 = 5; % x-coordinate of ending point
y2 = 7; % y-coordinate of ending point
dx = x2 - x1; % length of arrow in x-direction
dy = y2 - y1; % length of arrow in y-direction

figure; % create a new figure
hold on; % enable plot overlay

% plot the arrow
quiver(x1, y1, dx, dy, 0, 'linewidth', 2, 'maxheadsize', 0.8);

% add labels to the plot
xlabel('x');
ylabel('y');
title(


x1 = 1; % x-coordinate of starting point
y1 = 2; % y-coordinate of starting point
x2 = 5; % x-coordinate of ending point
y2 = 7; % y-coordinate of ending point
dx = x2 - x1; % length of arrow in x-direction
dy = y2 - y1; % length of arrow in y-direction

figure; % create a new figure
hold on; % enable plot overlay

% plot the arrow
quiver(x1, y1, dx, dy, 0, 'linewidth', 2, 'maxheadsize', 0.8);

% add labels to the plot
xlabel('x');
ylabel('y');
title('Arrow from (1,2) to (5,7)');

theta = linspace(0,2*pi,100);
radius = 2; % set the radius of the circle
x = radius*cos(theta);
y = radius*sin(theta);
plot(x,y)





% define circle
r = 1; % radius
c = [2, 0]; % center
t = linspace(0, 2*pi, 100);
x = c(1) + r*cos(t);
y = c(2) + r*sin(t);

% plot circle
figure;
h = plot(x, y);

% plot points with delay
for i = 1:5
    for j = 1:5
        pause(1); % pause for 1 second
        delete(h); % delete previous plot
        xj = c(1) + j - 1; % calculate x coordinate
        yi = c(2) + i - 1; % calculate y coordinate
        hold on;
        h = plot(xj, yi, 'ro'); % plot new point
        plot(x, y); % plot circle
        hold off;
        axis equal;
        xlim([c(1)-r-1, c(1)+r+1]); % set x limits to show entire circle
        ylim([c(2)-r-1, c(2)+r+1]); % set y limits to show entire circle
        drawnow;
    end
end
