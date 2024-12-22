% symbolic variables
syms the1 the2 the3 the4 the5 the6
syms a1 a2 a3 a4 a5 a6

% transformation matrices
H01 = [0, -cos(the1), sin(the1), 0;
       0, -sin(the1), -cos(the1), 0;
       1,         0,          0, a1;
       0,         0,          0, 1];

H12 = [cos(the2), -sin(the2), 0, a2*cos(the2);
       sin(the2), cos(the2),  0, a2*sin(the2);
       0,         0,          1, 0;
       0,         0,          0, 1];

H23 = [cos(the3), -sin(the3), 0, a3*cos(the3);
       sin(the3), cos(the3),  0, a3*sin(the3);
       0,         0,          1, 0;
       0,         0,          0, 1];

H34 = [0, -sin(the4), cos(the4), 0;
       0, cos(the4), sin(the4)  0;
       -1,         0,          0, a4;
       0,         0,          0, 1];

H45 = [cos(the5), 0, sin(the5), 0;
       sin(the5), 0, -cos(the5),  0;
       0,         1,          0, a5;
       0,         0,          0, 1];

H56 = [cos(the6), -sin(the6), 0, 0;
       sin(the6), cos(the6),  0, 0;
       0,         0,          1, a6;
       0,         0,          0, 1];
% Total transformation matrix
H06 = simplify(H01 * H12 * H23 * H34 * H45 * H56);

% Extract Px, Py, Pz from H05
Px = H06(1, 4);
Py = H06(2, 4);
Pz = H06(3, 4);

% Defining numerical values
a1_v = 199.34; a2_v = 250; a3_v = 250; a4_v = 109.1; 
a5_v = 108; a6_v = 75.86; pi=(22/7);
t1 = ((88.284+180)/180)*pi; 
t2 = ((-24.219+90)/180)*pi; 
t3 = (-113.870/180)*pi; 
t4 = ((-82.529+90)/180)*pi; 
t5 = ((-90+13.887)/180)*pi; 
t6 = (38.496/180)*pi;

% Substituting values and compute Px, Py, Pz
px_new = vpa(subs(Px, [the1, the2, the3, the4, the5, the6, a1, a2, a3, a4, a5, a6], ...
               [t1, t2, t3, t4, t5, t6, a1_v, a2_v, a3_v, a4_v, a5_v, a6_v]));

py_new = vpa(subs(Py, [the1, the2, the3, the4, the5, the6, a1, a2, a3, a4, a5, a6], ...
               [t1, t2, t3, t4, t5, t6, a1_v, a2_v, a3_v, a4_v, a5_v, a6_v]));

pz_new = vpa(subs(Pz, [the1, the2, the3, the4, the5, the6, a1, a2, a3, a4, a5, a6], ...
               [t1, t2, t3, t4, t5, t6, a1_v, a2_v, a3_v, a4_v, a5_v, a6_v]));

% Display results
px_new
py_new
pz_new